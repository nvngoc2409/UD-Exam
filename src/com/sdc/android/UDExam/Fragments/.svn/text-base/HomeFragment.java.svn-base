package com.sdc.android.UDExam.Fragments;

import com.sdc.android.UDExam.Swipeytabs.R;
import com.sdc.android.UDExam.Swipeytabs.R.id;

import android.os.Bundle;
import android.support.v4.app.Fragment;
import android.support.v4.view.ViewPager;
import android.view.LayoutInflater;
import android.view.View;
import android.view.View.OnClickListener;
import android.view.ViewGroup;
import android.widget.Button;

public class HomeFragment extends Fragment implements OnClickListener{
	private static ViewPager _mViewPager;
	private Button bt_personal_test, bt_group_test, bt_advanced_test, bt_review, bt_friends, bt_help, bt_favourite, bt_history;
	public static Fragment init(ViewPager mViewPager) {
		_mViewPager = mViewPager;
		return new HomeFragment();
	}

	@Override
    public View onCreateView(LayoutInflater inflater, ViewGroup container, Bundle savedInstanceState) {
        ViewGroup root = (ViewGroup) inflater.inflate(R.layout.home, null);
        bt_personal_test = (Button) root.findViewById(id.bt_personal_test);
        bt_personal_test.setOnClickListener(this);
        bt_group_test = (Button) root.findViewById(id.bt_group_test);
        bt_group_test.setOnClickListener(this);
        bt_advanced_test = (Button) root.findViewById(id.bt_advanced_test);
        bt_advanced_test.setOnClickListener(this);
        bt_review = (Button) root.findViewById(id.bt_review);
        bt_review.setOnClickListener(this);
        bt_friends = (Button) root.findViewById(id.bt_friends);
        bt_friends.setOnClickListener(this);
        bt_help = (Button) root.findViewById(id.bt_help);
        bt_help.setOnClickListener(this);
        bt_favourite = (Button) root.findViewById(id.bt_favourite);
        bt_favourite.setOnClickListener(this);
        bt_history = (Button) root.findViewById(id.bt_history);
        bt_history.setOnClickListener(this);
        return root;
	}

	@Override
	public void onClick(View v) {
		if(v.getId() == id.bt_review){
			_mViewPager.setCurrentItem(1);
		}
		if(v.getId() == id.bt_personal_test){
			_mViewPager.setCurrentItem(2);
		}
		if(v.getId() == id.bt_group_test){
			_mViewPager.setCurrentItem(3);
		}
		if(v.getId() == id.bt_advanced_test){
			_mViewPager.setCurrentItem(4);
		}
		if(v.getId() == id.bt_history){
			_mViewPager.setCurrentItem(5);
		}
		if(v.getId() == id.bt_favourite){
			_mViewPager.setCurrentItem(6);
		}
		if(v.getId() == id.bt_friends){
			_mViewPager.setCurrentItem(7);
		}
		if(v.getId() == id.bt_help){
			_mViewPager.setCurrentItem(8);
		}
	}
}
